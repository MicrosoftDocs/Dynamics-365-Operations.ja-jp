---
title: Inventory Visibility の在庫配賦
description: この記事では、在庫配賦機能の設定方法と使用方法について説明します。これにより、専用の在庫を確保して、最も収益性の高いチャネルや顧客を確実に満たすことができます。
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762675"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibility の在庫配賦

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>ビジネス バックグラウンドと目的

多くの場合、組織は、最も重要な販売チャネル、顧客グループ、地域、およびプロモーション イベントに手持在庫を事前に割り当て、事前に割り当てられた在庫が他の使用から保護され、割り当てに関連する販売トランザクションでのみ使用できるようにする必要があります。 Inventory Visibility の在庫配賦は、販売運用計画プロセスのコンポーネントであり、実際の販売活動が発生、または販売注文が作成される前に行われます。

たとえば、Contoso という名前の会社が、人気のある自転車を生産しています。 残念ながら、最近のサプライ チェーンの混乱が、その自転車のすべての輸送中の在庫に影響を与えているため、Contoso の手持在庫は限られており、最大限に活用する必要があります。 Contoso は、オンライン販売と店頭販売の両方を行っています。 各販売チャネルには、会社の重要な企業パートナー (マーケットプレースおよび大手小売業者) が数社あり、企業パートナーは自転車の販売可能在庫の一部を自分たちのために確保することを求めています。 そのため、自転車会社は、チャネル間での在庫配分のバランスをとり、VIP パートナーの期待も管理する必要があります。 両方の目標を達成する最善の方法は、各チャンネルおよび小売業者が後で消費者に販売できる特定の配賦数量を受け取ることができるように、在庫配賦を使用することです。

在庫配賦には 2 つの基本的なビジネス目的があります:

- **在庫保護 (リング フェンシング)** – 組織は、優先順位付けされたチャネル、地域、VIP 顧客、子会社に、制限または限定された在庫を事前に割り当てます。 Inventory Visibility の配賦機能は、他の配賦、引当、その他の販売需要が、以前に割り当てた在庫に影響を与えないように、配賦在庫を保護することを目的としています。
- **過剰販売管理** – Inventory Visibility の配賦機能は、仮引当に基づく実際の販売トランザクションが有効な場合に、受領当事者 (例えば、チャネルや顧客グループ) が過剰消費しないように、以前の配賦数量に制限を設定することを目的としています。

## <a name="allocation-definition-in-inventory-visibility-service"></a>Inventory Visibility サービスの配賦定義

### <a name="allocation-virtual-pool"></a>割り当て仮想プール

Inventory Visibility の配賦機能では、現物在庫の数量は確保されませんが、使用可能な現物在庫の数量を参照して、初期の *割り当て可能な* 仮想プール数量を定義します。 Inventory Visibility の在庫配賦はソフト配賦です。 実際の販売トランザクションが発生する前に行われ、販売注文に依存しません。 たとえば、最終顧客が販売チャネルまたは小売店舗を訪れて購入する前に、最も重要な販売チャネルまたは大企業の小売業者に在庫を割り当てることができます。

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>在庫配賦と仮引当の違い

[仮引当](inventory-visibility-reservations.md) は通常、実際の販売トランザクション (販売注文明細行) にリンクされます。 配賦と仮引当の両方を個別に使用できますが、一緒に使用する場合は、割り当て後に仮引当を行う必要があります。 割り当てに対するほぼリアルタイムの消費を実現するために、まず在庫配賦を行い、次に配賦数量に対して仮引当を行うことをお勧めします。 詳細については、[仮引当として消費](#consume-to-soft-reserved) を参照してください。

在庫配賦機能を使用すると、販売プランナーや主要アカウント マネージャーが、配賦グループ (チャネル、地域、顧客グループなど) 間で重要な在庫を管理および事前配賦できます。 また、配賦数量に対する消費のリアルタイムの追跡、調整、および分析をサポートしているため、補充または再配賦を時間どおりに行うことができるようにします。 この機能は、配賦、消費、配賦残高をリアルタイムで把握できるため、即売会や販促イベントなどで特に重要です。

## <a name="terminology"></a>用語

在庫配賦の説明で役に立つ用語と概念を次に示します:

- **配賦グループ** – 販売チャネル、顧客グループ、注文タイプなど、配賦を所有するグループ。
- **配賦グループ値** – 各配賦グループの値。 たとえば、*Web* または *店舗* が販売チャネル配賦グループの値であるのに対し、*VIP* または *標準* が顧客配賦グループの値である場合があります。
- **配賦階層** – 配賦グループを階層的に結合する手段。 たとえば、*チャネル* を階層レベル 1、*地域* をレベル 2、*顧客グループ* をレベル 3 として定義できます。 在庫配賦時に、配賦グループの値を指定する際は、配賦階層の順序に従う必要があります。 たとえば、*Web* チャネル、*ロンドン* 地域、および *VIP* 顧客グループに 200 台の赤い自転車を割り当てることができます。
- **配賦可能** – 今後の配賦に使用できる数量を示す *仮想共通プール*。 これは、独自の式を使用して自由に定義できる計算メジャーです。 仮引当機能も使用している場合は、同じ式を使用して、配賦可能数量と引当可能数量を計算することをお勧めします。
- **配賦済** – 配賦グループにより使用可能な割り当てられたクォータを示す現物メジャー。 消費数量が追加されるのと同時に差し引かれます。
- **消費済** – 元の割当数量に対して消費された数量を示す現物メジャー。 この現物メジャーに数値が追加されると、割り当てられた現物メジャーは自動的に削減されます。

次の図は、在庫配賦のビジネス ワークフローを示しています。

![Inventory Visibility の配賦ビジネス ワークフロー。](media/inventory-visibility-allocation-flow.png "Inventory Visibility の配賦ビジネス ワークフロー。")

次の図は、配賦階層と配賦グループを示しています。 ここに示す *仮想共通プール* は、割り当て可能な数量です。

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title="Inventory Visibility の配賦階層" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

## <a name="set-up-inventory-allocation"></a>在庫配賦の設定

在庫配賦機能は、次のコンポーネントで構成されます:

- 事前に定義された配賦関連のデータ ソース、現物メジャー、および計算メジャー。
- 最大 8 つのレベルを持つカスタマイズ可能な配賦グループ。
- 一連の配賦アプリケーション プログラミング インターフェイス (API):

    - 配賦
    - 再配賦
    - 未配賦
    - 消費
    - クエリ

配賦機能を構成するプロセスには、次の 3 つの手順があります:

- **構成 \> 機能管理と設定 \> 配賦** に移動して、Inventory Visibility アプリの機能を有効にします。
- [データ ソース](inventory-visibility-configuration.md#data-source-configuration) とその [メジャー](inventory-visibility-configuration.md#data-source-configuration-physical-measures) を設定します。
- 配賦グループの名前と階層を設定します。

### <a name="predefined-data-source"></a>事前定義済データ ソース

配賦機能を有効にして構成の更新 API を呼び出す場合、Inventory Visibility は、1 つの事前定義済データ ソースと複数の初期メジャーを作成します。

データ ソースは `@iv` という名前です。 既定の現物メジャーのセットが含まれます。 **構成 \> データ ソース** に移動して、Inventory Visibility アプリから表示できます。 **Datasource - @IV** が表示されます。 `@iv` データ ソースを展開して、初期現物メジャーの一覧を表示します:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

**計算メジャー** タブを選択して、`@iv.@available_to_allocate` という名前の初期の計算メジャーを表示します:

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>他の現物メジャーへの配賦可能数量の計算メジャーの追加

配賦を使用するには、割り当て可能な計算メジャー (`@iv.@available_to_allocate`) の式を正しく設定する必要があります。 たとえば、`fno` データ ソースと `onordered` メジャー、および `pos` データ ソースと `inbound` メジャーがあり、`fno.onordered` と `pos.inbound` の合計に対して手持在庫で割り当てを行うとします。 この場合、`@iv.@available_to_allocate` には、式に `pos.inbound` と `fno.onordered` を含める必要があります。 次に例を示します:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> データ ソース `@iv` は、定義済みのデータ ソースであり、接頭語 `@` 付きの `@iv` で定義された物理メジャーは事前に定義されたメジャーです。 これらのメジャーは配賦機能の事前に定義された構成なので、配賦機能を変更または削除したり、配賦機能を使用するときに予期しないエラーが発生する可能性があります。
>
> 定義済の計算メジャー `@iv.@available_to_allocate` に新しい物理メジャーを追加できますが、名前は変更してはなりません。

### <a name="manage-allocation-groups"></a>配賦グループの管理

最大で 8 つの配賦グループ名を設定できます。 グループには階層があります。 配賦グループを表示および更新するには、次の手順に従います。

1. Power Apps 環境にサインインし、**Inventory Visibility** を開きます。
1. **構成** ページを開き、**配賦** タブで **構成の編集** を選択します。 既定では、次の 4 つのレイヤーを持つ配賦階層があります: `Channel` (トップ レイヤー)、`customerGroup` (2 番目のレイヤー)、`Region` (3 番目のレイヤー)、`OrderType` (4 番目のレイヤー)。
1. 既存の配賦グループを削除するには、その横の **X** を選択します。 階層に新しい配賦グループを追加するには、新しい各グループの名前をフィールドに直接入力します。

    > [!IMPORTANT]
    > 配賦階層マッピングを削除または変更する場合は注意が必要です。 ガイダンスについては、[配賦の使用に関するヒント](#allocation-tips) を参照してください。

1. 配賦グループと階層設定の構成が完了したら、変更を保存し、右上の **構成の更新** を選択します。 構成済配賦グループの値は、ユーザー インターフェイスまたは API POST (/api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation/<wbr>allocate) を使用して配賦を作成すると更新されます。 両方のアプローチの詳細については、この記事の後半で説明します。

4 つのグループ名を使用し、\[`channel`、`customerGroup`、`region`、`orderType`\] に設定した場合、これらの名前は、構成の更新 API を呼び出す際に配賦関連の要求に対して有効になります。

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a>配賦の使用に関するヒント

- すべての製品について、配賦機能は、[製品インデックス階層の構成](inventory-visibility-configuration.md#index-configuration) で設定した製品インデックス階層に従って同じ *分析コード レベル* で使用する必要があります。 たとえば、インデックス階層が \[`Site`、`Location`、`Color`、`Size`\] であるとします。 分析コード レベル \[`Site`、`Location`、`Color`\] で 1 つの製品に対してある数量を割り当てる場合は、次回この製品を割り当てるときに同じレベル \[`Site`、`Location`、`Color`\] で割り当てる必要があります。 レベル \[`Site`、`Location`、`Color`、`Size`\] または \[`Site`、`Location`\] を使用すると、データに一貫性がなくなります。
- **配賦グループと階層の変更:** システムに配賦データが既に存在する場合、既存の配賦グループの削除や、配賦グループ階層のシフトにより、配賦グループ間の既存のマッピングが損なわれます。 そのため、新しい構成を更新する前に、古いデータはすべて手動でクリーンアップしてください。 ただし、最下位の階層に新しい配賦グループを追加しても既存のマッピングには影響しないので、データをクリーンアップする必要はありません。
- 配賦は、製品にプラスの `available_to_allocate` 数量がある場合にのみ成功します。
- 高 *配賦レベル* のグループからサブグループに製品を割り当てるには、`Reallocate` API を使用します。 たとえば、配賦グループ階層 \[`channel`、`customerGroup`、`region`、`orderType`\] があり、一部の製品を配賦グループ \[Online、VIP\] からサブ配賦グループ \[Online、VIP、EU\] に割り当てる場合は、`Reallocate` API を使用して数量を移動します。 `Allocate` API を使用すると、仮想共通プールから数量が割り当てられます。
- 製品の全体的な在庫状態 (共通プール) を表示するには、[手持在庫をクエリする](inventory-visibility-api.md#query-on-hand) API を使用して、*割り当て可能* な在庫金額を要求します。 その後、この情報に基づいて配賦決定を行います。

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a>配賦 API を使用する

現在、5 つの配賦 API が公開されています:

- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate** – この API を使用して初期割り当てを作成します。
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/unallocate** – この API を使用して、配賦数量を元に戻したり削除したりします。
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/reallocate** – この API を使用して、配賦数量を既存の配賦から他の配賦グループに移動します。
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/consume** – この API を使用して、配賦数量を差し引きます (使用します)。
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/query** – この API を使用して、既存の配賦レコードを配賦グループおよび階層と照合します。

### <a name="allocate"></a>配賦

`Allocate` APIを呼び出して、特定の分析コードを持つ製品を割り当てます。 要求本文のスキーマを次に示します。

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

たとえば、製品 *自転車*、サイト *1*、場所 *11*、色 *赤*、チャネル *オンライン*、顧客グループ *VIP*、地域 *米国* に対して、数量 10 を割り当てるとします。 この割り当てを行うには、次の本文内容を含む呼び出しを行うことができます。

```json
{
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

値は常に 0 (ゼロ) より大きい必要があります。

### <a name="unallocate"></a>未配賦

`Unallocate` API を使用して `Allocate` 操作を取り消します。 `Allocate` 操作では、負の数量は使用できません。 `Unallocate`の本文は `Allocate` の本文と同じです。

### <a name="reallocate"></a>再配賦

一部の配賦数量を別のグループの組み合わせに移動するには、`Reallocate` API を使用します。 要求本文のスキーマを次に示します。

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "groups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

たとえば、`Reallocate` API を呼び出して次の本文テキストを指定することで、分析コード \[site=1、location=11、color=red\] を持つ 2 台の自転車を配賦グループ \[Online、VIP、US\] から配賦グループ \[Online、VIP、EU\] に移動できます。

```json
{
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

### <a name="consume"></a>消費

`Consume` API を使用して、配賦に対する消費数量を転記します。 たとえば、この API を使用して、複数の実際のメジャーに移動できます。 要求本文のスキーマを次に示します。

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

たとえば、配賦グループ \[Online、VIP、US\] に分析コード \[site=1、location=11、color=red\] を持つ 8 台の割り当て済み自転車があるとします。 次の配賦可能数量の式が使用されます:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

8 台の自転車が `pos.inbound` メジャーから割り当てられます。

これで、3 台の自転車が販売され、配賦プールから取り出されます。 この移動を登録するには、次の要求本文を含む呼び出しを行うことができます。

```json
{
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

この呼び出し後、製品の配賦数量は 3 減少します。 さらに、Inventory Visibility は、`pos.inbound` = *-3* の手持在庫変更のイベントを生成します。 または、`pos.inbound` 値を維持し、配賦数量だけを消費することもできます。 ただし、この場合、消費数量を維持するために別の現物メジャーを作成するか、事前定義済メジャー `@iv.@consumed` を使用する必要があります。

この要求では、comsume 要求本文で使用する現物メジャーは、計算メジャーで使用されるモディファイア タイプに対して、反対のモディファイア タイプ (加算または減算) を使用する必要があります。 したがって、この consume 本文では、`iv.inbound` は 値 `Addition` ではなく `Subtraction` です。

Inventory Visibility が `fno` データ ソースのデータを変更できないことを常に主張したため、`fno` データ ソースを consume 本文で使用できません。 データ フローは一方向であるため、`fno` データ ソースに対するすべての数量変更は、Supply Chain Management 環境から取得される必要があります。

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>仮引当として消費

`Consume` API では、配賦数量を仮引当として消費することもできます。 この場合、`Consume` 操作は配賦数量を減らし、その数量に対して仮引当を行います。 この方法を使用するには、Inventory Visibility の [仮引当](inventory-visibility-reservations.md) 機能も使用する必要があります。

たとえば、仮引当現物メジャーを `iv.softreserved` として設定したとします。 次の式は、引当可能数量の計算メジャーに使用されます:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved`

配賦機能でこの設定を使用するには、`@iv.@allocated` を `iv.available_to_reserve` に追加して、次の式を生成します:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved` – `@iv.@allocated`

次に、`@iv.@available_to_allocate` を同じ値に更新します。

数量 3 を消費し、この数量を直接引当する場合は、次の要求本文を含む呼び出しを行うことができます。

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

この要求では、`iv.softreserved` 値が `Subtraction` ではなく `Addition` であることに注意してください。

### <a name="query"></a>クエリ

`Query` API を使用して、一部の製品の配賦関連情報を取得します。 分析コード フィルターおよび配賦グループ フィルターを使用して、結果を絞り込むことができます。 分析コードは、取得する分析コードと完全に一致する必要があります (たとえば、\[site=1、location=11\] は、\[site=1、location=11、color=red\] に対して関連性のない結果となります)。

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

たとえば、\[site=1、location=11、color=red\] グループと空のグループ フィールドを使用すると、すべての配賦レコードを取得できます:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

\[site=1、location=11、color=red\] とグループ \[channel=Online、customerGroup=VIP、region=US\] を使用すると、このグループの配賦レコードを取得できます:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>配賦ユーザー インターフェイスの使用

ユーザー インターフェイスを使用して配賦を手動で管理するには、Inventory Visibility アプリを開き、**運用可視化 \> 配賦** に移動します。 そこから、次のサブセクションで説明されているアクションを実行できます。

### <a name="create-an-allocation"></a>配賦の作成

次の手順に従って、Inventory Visibility アプリの **配賦** ページから配賦を作成します。

1. **配賦** を選択します。
1. 基本フィールド、分析コード、およびターゲット配賦グループの値を設定します。 **分析コード** セクションで collect データ ソースを選択したら、最初にドロップダウン リストを使用して分析コードを指定します (例: `siteId`)。 次に、表示されるフィールドに分析コード値を入力します。)
1. **送信** を選択します。

### <a name="consume-an-allocation"></a>配賦の消費

**消費** を選択して配賦を消費します。 適切な配賦グループと階層内で確実に消費を行うには、配賦の作成時に入力したのと同じ組織と分析コードの詳細のセットを入力します。

### <a name="reallocate-an-allocation"></a>配賦の再配賦

**再配賦** を選択して、既存の配賦数量を配賦グループのセットから別のセットに移動します。

### <a name="query-existing-allocations"></a>既存配賦のクエリ

**クエリ** を選択し、製品、組織、分析コード、および配賦グループの値を入力して、既存の配賦のクエリの結果を取得します。
