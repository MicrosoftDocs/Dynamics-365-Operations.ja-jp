---
title: Inventory Visibility の予約
description: この記事では、Inventory Visibility を使用して、引当を作成したり、引当を消費したり、指定された在庫量の引当を解除するために引当機能を設定する方法について説明します。
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
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762744"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility の予約

[!include [banner](../includes/banner.md)]

この記事では、仮引当の一般的なユース ケースについてと、Inventory Visibility での設定方法について説明します。 これには、仮引当の作成方法、物理的に消費する際にオフセットする方法、指定した在庫数量の調整や引当解除する方法に関する情報も含まれます。

## <a name="sample-use-case-for-soft-reservation"></a>仮引当のユース ケースの例

仮引当を使用すると、組織は利用可能な在庫に対する単一の確実なソース (特に注文のフルフィルメント プロセス中) を達成することができます。 これは、次の条件が存在する組織に便利な機能です。

- 組織に、出荷注文を直接処理する 2 つ以上のシステムがある。
- 組織は非常に厳格で、複数のシステムで起こりうる最後の在庫の重複予約を回避したい。 この状況は、すべての注文システムが Inventory Visibility に対して仮引当のインスタント API 呼び出しを行う場合に回避することができ、在庫の入手可能性を単一の確実なソースを入手できます。

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title="在庫可視化の仮引当" width="720" />](media/inventory-visibility-soft-reservation.png)

前の図は、仮引当の機能を表し、次の操作に焦点を当てています。

- 最初の在庫レベルは、Microsoft Dynamics 365 Supply Chain Management の Inventory Visibility に同期されています。
- 仮引当は、各注文のチャネルやシステムから Inventory Visibility に転記されます。 Inventory Visibility では、在庫状況が検証され、仮引当が実行されます。 仮引当に成功した場合、Inventory Visibility は仮引当済数量に追加され、引当可能 (AFR) 数量から控除されて、仮引当 ID を使用して応答します。
- この時点では、物理的な在庫数量は変わりません。
- その後、単一または集計された仮引当済注文 (注文行) を Supply Chain Management に同期して、確定引当を実行して倉庫にリリースするか、最終在庫数量を更新することができます。
- Supply Chain Management で物理的な在庫が更新されたときに [仮引当をオフセットする](#offset-scm) ようにシステムを設定できます。

通常は、Inventory Visibility サービスへの API 呼び出しを使用して、引当が作成、消費、およびキャンセルされます。

> [!NOTE]
> オプションで、Supply Chain Management (および他のサード パーティ システム) を設定して、Inventory Visibility を使用し、引当された数量を自動的にオフセットできます。 相殺数量は、Inventory Visibility の引当レコードから削除されます。
>
> 既定では、仮引当機能を有効にすると、オフセット機能が自動的に有効になります。

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>引当機能を有効にし設定する

引当機能を有効にするには、次の手順を実行します。

1. Power Apps にサインインして、**Inventory Visibility** を開きます。
1. **構成** ページを開きます。
1. **機能管理** タブで、*OnHandReservation* 機能を有効にします。
1. Supply Chain Management 環境にサインインします。
1. **[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ワークスペースに移動し、*引当相殺と Inventory Visibility の統合* 機能を有効にします (バージョン10.0.22 以降が必要)。
1. **在庫管理 \> 設定 \> Inventory Visibility 統合パラメーター** に移動し、**引当相殺** タブを開き、次の設定を行います。

    - **引当相殺を有効にする** – *はい* に設定し、この機能を有効にします。
    - **引当オフセット モディファイアー** – Inventory Visibility で行われた引当をオフセットする在庫トランザクションの状態を選択します。 この設定は、相殺をトリガーする注文処理ステージを決定します。 ステージは、注文の在庫トランザクション状態によって追跡されます。 次の値からいずれか 1 つを選択します。

        - *受注中* – 状態が *受注中* の注文は、作成されるとオフセット要求を送信します。 オフセット数量は作成された注文 (行) の数量になります。
        - *引当* – 状態が *引当* の注文は、注文の引当か物理的な引当かのいずれかの場合にオフセット要求を送信します。 *引当* 状態でオフセットすると、注文は、ピック済みの引当に最も近い新しい在庫状態 (ピック、梱包明細の転記済、請求済など) でオフセット要求を送信します。 この動作は、Supply Chain Management の引当をスキップして別の在庫状態に進む場合 (倉庫にリリースしてピックし梱包する場合など) でも発生します。 要求がトリガーされるのは 1 回のみです。 ピック時にトリガーされた場合、梱包明細の転記時にオフセットは複製されません。 オフセット数量は、オフセットがトリガーされたときの在庫トランザクション状態の数量と同じになります (つまり対応する注文行での、*引当済注文*/*引当現物*、またはそれ以降の状態)。

1. Inventory Visibility アプリにもう一度サインインして **構成** ページに移動し、**仮引当** タブで、既定の仮引当階層を確認します。 必要に応じて、新しい分析コードを階層に追加します。
1. **仮引当マッピングの設定** セクションで、既定の設定を表示します。 既定では、仮引当在庫数量は、データ ソース `iv` の `softreservephysical` 物理メジャーに対して記録されます。 *引当で使用可能* 計算メジャーは、`availabletoreserve` にマップされます。 `availabletoreserve` 計算メジャーを更新する場合は、**構成** ページに移動してから、**計算メジャー** タブで計算メジャーを展開および変更します。

詳細については、[Inventory Visibility のコンフィギュレーション](inventory-visibility-configuration.md)を参照してください。

> [!NOTE]
> 引当階層は、引当の際に指定する必要がある分析コードの順序を表します。 これは、インデックス階層が手持在庫クエリで機能するのと同じ方法で機能しますが、単独で使用することで、ユーザーは分析コードの詳細を指定して、より正確な引当を行うことができます。
>
> 仮引当階層には、コンポーネントとして `SiteId` および `LocationId` が含まれている必要がありますが、これは Inventory Visibility のパーティション構成を構築するためです。

引当の構成方法の詳細については、[引当構成](inventory-visibility-configuration.md#reservation-configuration)を参照してください。

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Inventory Visibility で引当機能を使用する

引当 API を呼び出すと、システムは指定した商品と数量の引当をマークします。

以下は、シナリオと API クエリ本文のサンプルです。 Contoso は、eコマースの Web サイトで製品 D0002 (キャビネット) を販売しています。 お客様が、Web サイトで小さな赤いキャビネットを注文しました。 Contoso は、次の分析コードを使用してこの注文の処理を決定しました。

- 組織 ID = usmf
- サイト = 1
- 倉庫 = 11
- 製品 = D0002
- 色 = 赤
- サイズ = S

Contoso は既に、独自の eコマース システムで、Inventory Visibility への API 接続を設定しています。 注文が入ったとき、システムは API 呼び出しをトリガーし、Inventory Visibility でキャビネットの仮引当を実行します。

### <a name="create-soft-reservations-using-the-reservation-api"></a>引当 API を使用した仮引当の作成

引当は、Inventory Visibility サービスで、`/api/environment/{environmentId}/onhand/reserve` のようなサービスの URL に POST リクエストを送信することで行われます。

引当の場合、要求本文には、組織 ID、製品 ID、引当済数量、および分析コードが含まれている必要があります。

引当 API を呼び出す際に、要求本文のブール値 `ifCheckAvailForReserv` パラメーターを指定することで、引当の検証を制御できます。 `True` という値は検証が必要であることを意味するのに対し、`False` という値は検証が必要ないことを意味します。 既定値は [`True`] です。

引当をキャンセルしたり、指定した引当在庫数量を解除したい場合は、数量を負の値に設定し、`ifCheckAvailForReserv` パラメーターを `False` に設定して検証をスキップします。

以下は、前のコンテキストで販売注文を参照する要求本文の例です。

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

正常な仮引当要求は、各引当レコードの *仮引当 ID* を返します。 仮引当 ID は、個々の仮引当レコードの一意識別子ではなく、仮引当要求に関連付けられている製品 ID と分析コード値の組み合わせです。 正常な引当注文を Supply Chain Management か別の ERP システムに同期してオフセットを行う際に、注文ラインに仮引当 ID を記録できます。

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a>Supply Chain Management で仮引当をオフセットする

注文数量が Supply Chain Management か他の ERP システムで物理的に差し引かれる場合は、仮引当数量をオフセットできます。 Inventory Visibility で、Supply Chain Management と統合した仮引当オフセットを使用できるようになります。

仮引当をオフセットするには、次の手順に従います。

1. Supply Chain Management にサインインします。
1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. 外部販売注文をもう一度作成し、同じ製品 ID、組織、サイト、倉庫、および分析コード値を使用する販売ラインを追加します。
1. **販売注文明細行** FastTab で、入力した販売行を選択し、ツールバーで **在庫 \> 予約 ID** の順に選択します。
1. 次の手順のいずれかを実行します。

    - 仮引当要求の応答に仮引当 ID をコピーし、**引当 ID** フィールドに貼り付けます。
    - **予約 ID** を空白のままにし、**在庫可視化サービスの自動オフセット** チェックボックスをオンにします。 システムは、選択した行に入力された品目 ID および分析コード値に基づいて、オフセットする製品と製品分析コードを自動的に決定します。

1.  **OK** を選択します。
1. 同じ販売行を選択したまま、**販売注文行** FastTab のツールバーで **在庫 \> 引当** を選択して、注文数量を物理的に引き当てます。
1. 以前に **引当オフセット モディファイア―** フィールドを *引当済み* に設定した場合、注文行がの状態が *物理的な引当* か *引当注文* のときにオフセットがトリガーされます。 バッチ ジョブは 1 分に 1 回実行され、Supply Chain Management からのオフセット要求を Inventory Visibility に同期します。

> [!NOTE]
> 指定された引当オフセット モディファイアーを含むトランザクション状態は、次のすべての条件が満たされた場合に、トランザクションの更新により、対応する引当レコードがオフセットされます。
>
> - 在庫トランザクションでの引当 ID は、Inventory Visibility で引当レコードの引当 ID と一致します。
> - 在庫トランザクションの分析コードは、Inventory Visibility の引当レコードの分析コードと一致します。
> - 在庫トランザクション状態の変更は、在庫トランザクション状態が注文プロセスが完了またはスキップされたという事実を反映している場合に、引当に対する相殺をトリガーします。

オフセット数量は、関連する在庫トランザクションで指定された在庫数量に従います。 Inventory Visibility に引当済数量が残っている場合のみ、オフセットは有効になります。

### <a name="cancel-or-revert-a-soft-reservation"></a>仮引当をキャンセルまたは元に戻す

元の注文行がキャンセルまたは削除された場合に、対応する仮引当を元に戻す必要がある場合は、API クエリ本文にまったく同じ情報を含むマイナス数量を転記します。
