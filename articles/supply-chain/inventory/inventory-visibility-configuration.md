---
title: Inventory Visibility の構成
description: この記事では、Inventory Visibility を構成する方法について説明します。
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2a368535c9644e174d1a2460ac0891c9dc1b1b3f
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850026"
---
# <a name="configure-inventory-visibility"></a>Inventory Visibility の構成

[!include [banner](../includes/banner.md)]

この記事では、Power Apps で Inventory Visibility アプリを使用して Inventory Visibility を構成する方法を説明します。

## <a name="introduction"></a><a name="introduction"></a>概要

Inventory Visibility の使用を開始する前に、この記事の説明に従って、次の構成を完了する必要があります:

- [データ ソースの構成](#data-source-configuration)
- [パーティションの構成](#partition-configuration)
- [製品インデックス階層の構成](#index-configuration)
- [引当の構成 (オプション)](#reservation-configuration)
- [クエリ プリロード構成 (オプション)](#query-preload-configuration)
- [既定の構成サンプル](#default-configuration-sample)

## <a name="prerequisites"></a>前提条件

開始する前に、[Inventory Visibility のインストールと設定](inventory-visibility-setup.md)で示されているように、Inventory Visibility アドインのインストールと設定を行います。

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Inventory Visibility アプリの構成ページ

Power Apps で、[Inventory Visibility アプリ](inventory-visibility-power-platform.md) の **構成** ぺージで手持構成および仮引当構成の設定をサポートします。 アドインをインストールすると、既定の構成に Microsoft Dynamics 365 Supply Chain Management (`fno` データ ソース) からの値が含まれます。 既定の設定を確認できます。 また、業務要件や外部システムの在庫転記要件に基づき、複数のシステム間で在庫変更を転記、整理、クエリする方法を標準化するように構成を変更することができます。 この記事の残りのセクションでは、**構成** ページの各部分の使い方について説明します。

構成の完了後、必ずアプリ内の **構成の更新** を選択してください。

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Power Apps の機能管理で Inventory Visibility 機能を有効にする

Inventory Visibility アドインは、Power Apps のインストールにいくつかの新機能を追加します。 既定では、これらの機能は無効になっています。 これらを使用するには、**構成** ページを開き、**機能管理** タブで必要に応じて以下の機能を有効にします。

| 機能管理名 | Description |
|---|---|
| *OnHandReservation* | この機能では、Inventory Visibility を使用して、引当を作成したり、引当を消費したり、指定された在庫量の引当を解除することができます。 詳細については、[Inventory Visibility 引当](inventory-visibility-reservations.md) を参照してください。 |
| *OnHandMostSpecificBackgroundService* | この機能は、すべての分析コードと共に、製品の在庫集計を提供します。 在庫集計データは、Inventory Visibility から定期的に同期されます。 既定の同期頻度は 15 分に 1 回で、5 分ごとに高く設定できます。 詳細については、[在庫概要](inventory-visibility-power-platform.md#inventory-summary) を参照してください。 |
| *OnHandIndexQueryPreloadBackgroundService* | この機能は、コンフィギュレーション済の分析コードに基づいて、一連の在庫集計データを定期的にフェッチして格納します。 日常業務に関連し、倉庫管理プロセス (WMS) に対して有効な品目と互換性のある分析コードのみを含む在庫集計を提供します。 詳細については、[事前読み込みされたオンハンド クエリをオンにして構成する](#query-preload-configuration) と [ストリームラインされたオンライン クエリを事前読み込みする](inventory-visibility-power-platform.md#preload-streamlined-onhand-query) を参照してください。 |
| *OnhandChangeSchedule* | このオプション機能により、手持在庫変更スケジュールと、納期回答可能在庫 (ATP) 機能が有効になります。 詳細については、[Inventory Visibility の手持変更スケジュールと納期回答可能在庫](inventory-visibility-available-to-promise.md) を参照してください。 |
| *割り当て* | このオプション機能により、Inventory Visibility で在庫保護 (リング フェンシング) および過剰販売管理の機能を使用することができます。 詳細については、[Inventory Visibility の在庫配賦](inventory-visibility-allocation.md) を参照してください。 |
| *Inventory Visibility で在庫品目を有効化* | このオプション機能によって、Inventory Visibility が有効になり、倉庫管理プロセス (WMS) が有効な品目がサポートされます。 詳細については、[WMS 品目に対応した Inventory Visibility](inventory-visibility-whs-support.md) を参照してください。 |

> [!IMPORTANT]
> *OnHandIndexQueryPreloadBackserviceService* 機能または *OnHandMostSpecificBackgroundService* 機能両方ではなく、どちらかを使用することをお勧めします。 両方の機能を有効にすることで、パフォーマンスに影響を与えます。

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>サービス エンドポイントを検索する

Inventory Visibility サービスの正しいエンドポイントが分からない場合、Power Apps の **構成** ページを開き、右上隅の **サービス詳細の表示** を選択します。 ページに正しいサービス エンドポイントが表示されます。 また、[Lifecycle Services 環境に応じたエンドポイントの検索](inventory-visibility-api.md#endpoint-lcs) にある説明に従って、Microsoft Dynamics Lifecycle Services でエンドポイントを検索することもできます。

> [!NOTE]
> 間違ったエンドポイントを使用すると、Supply Chain Management が在庫可視性に同期するときに Inventory Visibility のインストールが失敗し、エラーが発生する可能性があります。 エンドポイントがわからない場合は、システム管理者に問い合わせてください。 エンドポイントの URL では、次の形式を使用します。
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>データ ソースの構成

各データ ソースは、データの取得元のシステムを表しています。 データ ソース名の例には、`fno` (Supply Chain Management 対応) および `pos` ("販売時点管理" の略) が含まれます。 既定では、Supply Chain Management が Inventory Visibility の既定のデータ ソース (`fno`) として設定されます。

> [!NOTE]
> `fno` データ ソースは Supply Chain Management 用に予約されています。 Inventory Visibility アドインが Supply Chain Management 環境と統合されている場合は、データソースの `fno` に関連する設定を削除しないことをお勧めします。

データ ソースを追加するには、次の手順に従います。

1. Power Apps 環境にサインインし、**Inventory Visibility** を開きます。
1. **構成** ページを開きます。
1. **データ ソース** タブで、**新しいデータ ソース** を選択してデータ ソースを追加します (`ecommerce` またはわかりやすいデータ ソース ID など)。

> [!NOTE]
> データ ソースを追加する場合、Inventory Visibility サービスの構成を更新する前に、データ ソースの名前、物理的測定、および分析コードのマッピングを検証してください。 **構成の更新** を選択した後は、これらの設定を変更することはできません。

データ ソースの構成には、次の部分が含まれています。

- 分析コード (分析コード マッピング)
- 物理的測定
- 計算メジャー

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>分析コード (分析コード マッピング)

分析コードを構成する目的は、分析コードの組み合わせに基づいて、イベントやクエリを投稿する複数のシステム統合を標準化することです。 Inventory Visibility は、データ ソースの分析コードからマッピングできるベース分析コードの一覧を提供します。 33 個の分析コードをマッピングに使用することができます。

- データ ソースの 1 つとして Supply Chain Management を使用している場合、Supply Chain Management の標準分析コードに 13 の分析コードが既定でマップされています。 他の 12 の分析コード (`inventDimension1` から `inventDimension12`) が Supply Chain Management のカスタム分析コードにもマッピングされます。 残りの 8 つの分析コード (`ExtendedDimension1` から `ExtendedDimension8`) は、外部データ ソースにマップできる拡張分析コードです。
- データ ソースの 1 つとして Supply Chain Management を使用しない場合、分析コードを自由にマップすることができます。 使用可能な分析コードの完全な一覧を次の表に示します。

> [!NOTE]
> Supply Chain Management を使用し、Supply Chain Management と Inventory Visibility 間で既定の分析コード マッピングを変更した場合、変更された分析コードはデータを同期しません。 そのため、分析コードが既定の分析コードの一覧に含まれておらず、外部データ ソースを使用している場合は、`ExtendedDimension1` から `ExtendedDimension8` を使用してマッピングすることをお勧めします。

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
> 前の表で表示されていた分析コード タイプは、参照専用です。 Inventory Visibility で定義する必要はありません。
>
> 在庫 (カスタム) 分析コードは、Supply Chain Management に対して引当されている場合があります。 その場合、代わりに拡張分析コードを使用できます。

外部システムは、RESTful API を介して Inventory Visibility にアクセスできます。 統合の場合、Inventory Visibility では *外部データ ソース* と、*外部分析コード* から *ベース分析コード* へのマッピングを構成できます。 分析コードのマッピング テーブルの例を次に示します。

| 外部分析コード | ベース分析コード |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

分析コード マッピングを構成することで、外部分析コードを直接 Inventory Visibility に送信できます。 次に、Inventory Visibility は外部分析コードをベース分析コードに自動的に変換します。

分析コード マッピングを追加するには、次の手順に従います。

1. Power Apps 環境にサインインし、**Inventory Visibility** を開きます。
1. **構成** ページを開きます。
1. **データ ソース** タブで、分析コード マッピングを行うデータ ソースを選択します。 次に、**分析コード マッピング** セクションで **追加** を選択して、分析コード マッピングを追加します。

    ![分析コード マッピングの追加](media/inventory-visibility-dimension-mapping.png "分析コード マッピングの追加")

1. **分析コード名** フィールドで、ソース分析コードを指定します。
1. **終了分析コード** フィールドで、マップする Inventory Visibility の分析コードを選択します。
1. **保存** を選択します。

たとえば、製品の色分析コードが含まれる `ecommerce` という名前のデータ ソースを既に作成している場合、 マッピングを行うには、最初に `ProductColor` を `ecommerce` データ ソースの **分析コード名** フィールドに追加してから、**終了基準分析コード** フィールドの `ColorId` を選択します。

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>物理的測定

データ ソースが在庫の変更を Inventory Visibility に転記する場合、*物理的測定* を使用してその変更を転記します。 物理的測定は数量を変更し、在庫状態を反映します。 必要に応じて、独自の物理的測定を定義することができます。 クエリは、物理的測定に基づくことがあります。

Inventory Visibility は、Supply Chain Management (`fno` データ ソース) にマップされている既定の物理的測定の一覧を提供します。 これら既定の物理的測定は、Supply Chain Management (**在庫管理 \> 照会およびレポート \> 手持在庫リスト**) の **手持在庫リスト** ページにある在庫トランザクションの状態から取得されます。 次の表に、物理的測定の例を示します。

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

1. Power Apps 環境にサインインし、**Inventory Visibility** を開きます。
1. **構成** ページを開きます。
1. **データ ソース** タブで、物理的測定を追加するデータ ソース (`ecommerce` データ ソースなど) を選択します。 次に、**物理的測定** セクションで **追加** を選択し、測定名 (たとえば、このデータ ソースの返品数量を Inventory Visibility に記録する場合は `Returned` など) を指定します。 変更を保存します。

### <a name="extended-dimensions"></a>拡張された分析コード

データ ソースで外部データ ソースを使用する顧客は、`InventOnHandChangeEventDimensionSet` クラスと `InventInventoryDataServiceBatchJobTask` クラスの [クラス拡張機能](../../fin-ops-core/dev-itpro/extensibility/class-extensions.md) を作成することで Dynamics 365 が提供する拡張機能の利点を利用できます。

拡張機能を作成して、`InventSum` テーブルにカスタム フィールドを追加するために、データベースと同期してください。 この記事の 分析コード を参照して、カスタム分析コードを Inventory の `BaseDimensions` で在庫の 8 つの拡張分析コードにマップすることができます。

> [!NOTE] 
> 拡張機能の作成の詳細については、[拡張機能のホーム ページ](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) を参照してください。

### <a name="calculated-measures"></a>計算メジャー

Inventory Visibility を使用して、在庫の物理的測定と *カスタム計算測定* の両方を照会できます。 計算メジャーは、物理的測定の組み合わせで構成されるカスタマイズされた計算式を提供します。 この機能により、追加または削除される一連の物理的測定を定義して、カスタマイズされた測定を作成できるようになります。

> [!IMPORTANT]
> 計算メジャーは、現物メジャーの構成です。 その式には、計算メジャーではなく、重複しない現物メジャーのみを含めることができます。

構成により、加算の修飾子または減算の修飾子を含む一連の計算メジャー フォーミュラを定義して、合計集計された出来高数量を取得できます。

カスタム計算測定を設定するには、次の手順に従います。

1. Power Apps 環境にサインインし、**Inventory Visibility** を開きます。
1. **構成** ページを開きます。
1. **計算測定** タブで **新しい計測** を選択し、計算された測定を追加します。
1. 新しい計算メジャーについて、次のフィールドを設定します。

    - **新しい計算メジャー名** – 計算メジャーの名前を入力します。
    - **データ ソース** – 新しい計算メジャーを含めるデータ ソースを選択します。 照会しているシステムはデータ ソースです。

1. **追加** を選択して、モディファイアーを新しい計算メジャーに追加します。
1. 新しいモディファイアー用に次のフィールドを設定します。

    - **モディファイアー** – モディファイアー タイプ (*加算* または *減算*) を選択します。
    - **データ ソース** – モディファイアー値を提供するメジャーが含まれるデータ ソースを選択します。
    - **メジャー** – モディファイア―の値を提供するメジャーの名前 (選択したデータ ソースから) を選択します。

1. ATP に必要なすべての修飾子を追加し、計算メジャーのフォーミュラが完了するまで、手順 5 から 6 を繰り返します。
1. **保存** を選択します。

たとえば、ファッション会社は、次の 3 つのデータ ソースを使用して運営しています。

- `pos` – 店舗のチャネルに対応します。
- `fno` – Supply Chain Management に対応します。
- `ecommerce` – Web チャネルに対応します。

サイト 1、倉庫 11、`ColorID` 分析コードの値が `Red` の製品 D0002 (キャビネット) にクエリを実行する場合、計算メジャーがないと、構成済の物理的測定ごとに在庫数量を表示するクエリ結果が次のようになります。 ただし、データ ソース全体の引当数量に対する利用可能な合計の可視性は確保できません。

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
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
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

この計算式を使用すると、新しいクエリ結果にカスタマイズされた測定が含まれます。

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

カスタム測定での計算設定に基づく `MyCustomAvailableforReservation` の出力は、100+50–10+80–20+90+30–60–40=220 となります。

## <a name="partition-configuration"></a><a name="partition-configuration"></a>パーティションの構成

現在、パーティション構成は、データの分散方法を示す 2 つの基本分析コード (`SiteId` と `LocationId`) で構成されています。 同じパーティションで運用することで、より高いパフォーマンスを低コストで実現できます。 次の表は、Inventory Visibility アドインが提供する規定のパーティション構成です。

| ベース分析コード | 階層 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

ソリューションには、このパーティション構成が規定で含まれています。 したがって、 *自分で定義する必要はありません*。

> [!IMPORTANT]
> 既定のパーティション構成をカスタマイズしないでください。 それを削除したり変更したりすると、予期せぬエラーが発生する可能性があります。

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>製品インデックス階層の構成

多くの場合、手持在庫クエリは、最高「合計」レベルのみだけではありません。 代わりに、在庫分析コードに基づいて集計される結果も表示することができます。

Inventory Visibility は、クエリのパフォーマンスを向上させるための *インデックス* を設定することで、柔軟性を高めることができます。 これらのインデックスは、分析コードまたは分析コードの組み合わせに基づいています。 インデックスは、次の表で定義されているように、*セット番号*、*分析コード*、および *階層* で構成されています。

| 氏名 | 説明 |
|---|---|
| セット番号 | 同じセット (インデックス) に属する分析コードはグループ化され、同じセット番号が割り当てされます。 |
| 分析コード | クエリ結果が集計されるベース分析コード。 |
| 階層 | この階層を利用して、フィルターやグループごとのクエリ パラメーターで使用する際に、特定のディメンションの組み合わせのパフォーマンスを向上させることができます。 たとえば、`(ColorId, SizeId, StyleId)` という階層順序でディメンション セットを設定すると、4 つのディメンションの組み合わせに関連するクエリをより迅速に処理することができます。 最初の組み合わせは空、2 番目が `(ColorId)`、3 番目が `(ColorId, SizeId)`、4 番目が `(ColorId, SizeId, StyleId)` です。 その他の組み合わせは高速化されません。 フィルターには順番の製薬はありませんが、性能を向上させる場合は、このディメンションの範囲内である必要があります。 詳細については、次の例を参照してください。 |

製品階層インデックスを設定するには、以下の手順に従ってください。

1. Power Apps 環境にサインインし、**Inventory Visibility** を開きます。
1. **構成** ページを開きます。
1. **製品階層インデックス** タブの **分析コード マッピング** セクションで **追加** を選択して、分析コード マッピングを追加します。
1. 既定では、インデックスの一覧が用意されています。 既存のインデックスを変更するには、関連するインデックスのセクションで **編集** または **追加** を選択します。 新しいインデックス セットを作成するには、**新しいインデックス セット** を選択します。 すべてのインデックス セットの各行の **分析コード** フィールドで、ベース分析コードの一覧から選択します。 次のフィールドの値は自動的に生成されます。

    - **セット番号** – 同じグループ (インデックス) に属する分析コードはグループ化され、同じセット番号が割り当てされます。
    - **階層** – 階層化により、フィルタやグループごとのクエリ パラメーターで使用する場合、特定のディメンションの組み合わせのパフォーマンスが向上します。

> [!TIP]
> インデックス階層を設定する際に注意が必要なヒントをいくつか示します:
>
> - パーティション構成で定義されたベース分析コードは、インデックス構成で定義しないでください。 基本分析コードがインデックス構成で再度定義された場合は、このインデックスでクエリすることはできません。
> - すべての分析コードの組み合わせによって集計された在庫のみをクエリする必要がある場合は、基本分析コード `Empty` を含む単一のインデックスを設定します。

### <a name="example"></a>例

このセクションでは、階層の仕組みを示す例を提供します。

次の表に、このサンプルで使用可能な在庫の一覧を示します。

| 品目 | ColorId | SizeId | StyleId | Quantity |
|---|---|---|---|---|
| D0002 | 黒 | 小 | ワイド | 1 |
| D0002 | 黒 | 小 | 通常 | 2 |
| D0002 | 黒 | 大 | ワイド | 3 |
| D0002 | 黒 | 大 | 通常 | 4 |
| D0002 | 赤 | 小 | ワイド | 5 |
| D0002 | 赤 | 小 | 通常 | 6 |
| D0002 | 赤 | 大 | 通常 | 7 |

インデックス階層の設定方法を次の表に示します。

| 設定番号 | 分析コード | 階層 |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

インデックスを使用すると、次の方法で手持在庫をクエリできます。

- `()` – すべてグループ化されます

    - D0002、28

- `(ColorId)` – `ColorId` 別にグループ化されます

    - D0002、黒、10
    - D0002、赤、18

- `(ColorId, SizeId)` – `ColorId` と `SizeId` の組み合わせ別にグループ化されます

    - D0002、黒、S、3
    - D0002、黒、L、7
    - D0002、赤、S、11
    - D0002、赤、L、7

- `(ColorId, SizeId, StyleId)` – `ColorId`、`SizeId` および `StyleId` の組み合わせ別にグループ化されます

    - D0002、黒、S、ワイド、1
    - D0002、黒、S、通常、2
    - D0002、黒、L、ワイド、3
    - D0002、黒、L、通常、4
    - D0002、赤、S、ワイド、5
    - D0002、赤、S、通常、6
    - D0002、赤、L、通常、7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>引当の構成 (オプション)

仮引当機能を使用する場合は、引当の構成が必要です。 構成は 2 つの基本的な部分で構成されています。

- 仮引当マッピング
- 仮引当階層

### <a name="soft-reservation-mapping"></a>仮引当マッピング

引当を行う際に、手持在庫が現在引当可能であるかどうかについて知りたい場合があります。 検証は、物理的測定の組み合わせの計算式を表す計算メジャーにリンクされます。

物理的測定から計算メジャーへのマッピングを設定することにより、Inventory Visibility サービスを有効にし、物理的測定に基づいて、引当可能在庫数を自動的に検証することができます。

このマッピングを設定する前に、(この記事で前述されているように) Power Apps の **構成** ページの **データ ソース** タブと **計算メジャー** タブで、現物メジャー、計算メジャー、およびそれらのデータ ソースを定義する必要があります。

仮引当マッピングを定義するには、次の手順に従います。

1. 仮引当測定として機能する物理的測定を定義します (`SoftReservPhysical` など)。
1. **構成** ページの **計算メジャー** タブで、物理的計測にマップする AFR 計算式を含む、*引当に使用可能な* (AFR) 計算メジャーを定義します。 たとえば、`AvailableToReserve` (引当に使用可能) を設定し、以前に定義された `SoftReservPhysical` 物理的測定にマップすることができます。 このようにして、引当に使用可能になる `SoftReservPhysical` 在庫状態の数量を検索できます。 次の表は、AFR 計算式を示しています。

    | 計算タイプ | データ ソース | 物理的測定 |
    |---|---|---|
    | 加算 | `fno` | `AvailPhysical` |
    | 加算 | `pos` | `Inbound` |
    | 減算 | `pos` | `Outbound` |
    | 減算 | `iv` | `SoftReservPhysical` |

    引当測定の基になる物理的測定が含まれるように、計算メジャーを設定することをお勧めします。 このようにして、計算メジャー数量は、引当測定数量の影響を受けます。 したがって、この例では、`iv` データー ソースの `AvailableToReserve` 計算メジャーには、コンポーネント として `iv` からの `SoftReservPhysical` 物理測定を含む必要があります。

1. **構成** ページを開きます。
1. **仮引当マッピング** タブで、物理的測定から計算メジャーへのマッピングを設定します。 前の例の場合、次の設定を使用して、以前に定義された `SoftReservPhysical` 物理測定に `AvailableToReserve` をマップすることができます。

    | 物理的測定データ ソース | 物理的測定 | 引当データ ソースで使用可能 | 引当計算メジャーで使用可能 |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > **仮引当マッピング** タブで編集できない場合、**機能管理** タブの *OnHandReservation* 機能を有効にしなければならない場合があります。

これで、`SoftReservPhysical` で引当を行うと、Inventory Visibility によって自動的に `AvailableToReserve` とその関連計算式が検出され、引当の検証が行われます。

たとえば、Inventory Visibility に次の手持在庫があるとします。

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservPhysical`  
=70+50–20–90  
=10

したがって、`iv.SoftReservPhysical` で引当を行う場合、数量が `AvailableToReserve` (10) 以下であれば、仮引当要求に成功します。

> [!NOTE]
> 引当 API を呼び出す際に、要求本文のブール値 `ifCheckAvailForReserv` パラメーターを指定することで、引当の検証を制御できます。 `True` は検証が必要であることを表し、`False` は検証が必要でないことを表します (`AvailableToReserve` の結果数量がマイナスの場合でも、仮引当を実行できます)。 既定値は [`True`] です。

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

## <a name="available-to-promise-configuration-optional"></a>納期回答可能在庫の構成 (オプション)

Inventory Visibility を設定すると、今後の手持在庫変更をスケジュールし、納期回答可能在庫 (ATP) 数量を計算できます。 ATP は、使用可能な品目の数量で、次の期間に顧客に約束できます。 この計算を使用すると、注文のフルフィルメント機能を大幅に強化できます。 この機能を使用するには、**機能管理** タブでこの機能を有効にして、**ATP 設定** タブで設定する必要があります。詳細については、[Inventory Visibility の手持在庫変更スケジュールおよび納期回答可能在庫](inventory-visibility-available-to-promise.md) を参照してください。

## <a name="turn-on-and-configure-preloaded-on-hand-queries-optional"></a><a name="query-preload-configuration"></a>事前読み込みされたオンハンド クエリをオンにして構成する (オプション)

在庫可視化は、事前構成済みの分析コードに基づいて、一連の在庫集計データを定期的にフェッチして格納します。 これには次のメリットがあります。

- 日次業務に関連する分析コードのみを含む在庫集計を格納する項目ビュー。
- 倉庫管理プロセス (WMS) に対して有効な品目と互換性のある在庫集計。

設定後にこの機能を使用 する方法の詳細については、[合理化されたオンハンド クエリを事前に読み込む](inventory-visibility-power-platform.md#preload-streamlined-onhand-query) を参照してください。

> [!IMPORTANT]
> *OnHandIndexQueryPreloadBackserviceService* 機能または *OnHandMostSpecificBackgroundService* 機能両方ではなく、どちらかを使用することをお勧めします。 両方の機能を有効にすることで、パフォーマンスに影響を与えます。

これらの手順に従って、機能を設定します。

1. 在庫可視化 Power App にサインインします。
1. **構成 \> 機能管理と設定** の順に移動します。
1. *OnHandIndexQueryPreloadBackqueryservice* 機能が既に有効になっている場合は、クリーンアップ プロセスの完了に非常に長い時間がかかる可能性があるから、この機能をオフにすることをお勧めします。 この手順の後半で、それをサイドオンにします。
1. **事前読み込み設定** タブを開きます。
1. **手順 1: 事前読み込みストレージのクリーンアップ** セクションで、**クリーンアップ** を選択してデータベースをクリーンアップし、新しいグループ化の設定を受け入れる準備をします。
1. **手順 2: グループ結果のグループ化** セクションの **結果を以下でグループ化** フィールドに、クエリ結果をグループ化するフィールド名のコンマ区切り一覧を入力します。 事前読み込みストレージ データベースにデータが格納された後は、前の手順の説明に従ってデータベースをクリーンアップするまで、この設定を変更できません。
1. **構成 \> 機能管理と設定** の順に移動します。
1. *OnHandIndexQueryPreloadBackgroundService* 機能をオンにします。
1. 変更をコミットするには、**構成** の右上隅にある **構成の更新** を選択します。

## <a name="complete-and-update-the-configuration"></a>構成の完了と更新

構成が完了した後、すべての変更を Inventory Visibility にコミットする必要があります。 これらの手順に従って変更します。

1. Power Apps の **構成** ページで、右上隅にある **構成の更新** を選択します。 
1. システムは、サインイン資格情報を要求します。 次の値を入力します。

    - **クライアント ID** – Inventory Visibility のために作成した Azure アプリケーション ID。
    - **テナント ID** – Azure テナント ID。
    - **クライアント シークレット** – Inventory Visibility のために作成した Azure アプリケーション シークレット。

    これらの資格情報の詳細については、[Inventory Visibility のインストールと設定](inventory-visibility-setup.md) を参照してください。

    > [!IMPORTANT]
    > 構成を更新する前に、データ ソースの名前、物理的測定、および分析コードのマッピングを検証してください。 更新した後は、これらの設定を変更することはできません。

1. サインイン後、**構成の更新** を再度選択します。 設定が適用され、変更された内容が表示されます。

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>既定の構成サンプル

初期化の段階では、Inventory Visibility が既定の構成を設定しますが、その詳細はこちらをごらんください。 必要に応じてこの構成を変更できます。

### <a name="data-source-configuration"></a>データ ソースの構成

#### <a name="configuration-of-the-iv-data-source"></a>iv データ ソースの構成

このセクションでは、`iv` データ ソースの構成方法について説明します。

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>"iv" データ ソース用に構成された現物メジャー

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
| 追加 | `fno` | `ReservPhysical` |
| 追加 | `fno` | `ReservOrdered` |
| 追加 | `iv` | `ReservPhysical` |
| 追加 | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>"fno" データ ソースの構成

このセクションでは、`fno` データ ソースの構成方法について説明します。

##### <a name="dimension-mappings-for-the-fno-data-source"></a>"fno" データ ソースの分析コード マッピング

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

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>"fno" データ ソース用に構成された現物メジャー

次の物理的測定は、`fno` データ ソース用に構成されています。

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

#### <a name="configuration-of-the-pos-data-source"></a>"pos" データ ソースの構成

このセクションでは、データ ソース `pos` の構成方法について説明します。

##### <a name="physical-measures-for-the-pos-data-source"></a>"pos" データ ソース用の現物メジャー

次の物理的測定は、`pos` データ ソース用に構成されています。

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity 計算メジャー

次の表に示すように、`AvailQuantity` 計算メジャーは `pos` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 追加 | `fno` | `AvailPhysical` |
| 追加 | `pos` | `PosInbound` |
| 減算 | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>"iom" データ ソースの構成

次の物理的測定は、`iom` (Intelligent Order Management) データ ソース用に構成されています。

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>"erp" データ ソースの構成

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
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>引当階層

次の表に、既定の引当階層を示します。

| ベース分析コード | 階層 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
