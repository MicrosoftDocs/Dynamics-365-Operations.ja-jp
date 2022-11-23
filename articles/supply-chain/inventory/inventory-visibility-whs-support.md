---
title: WMS 品目に対応した Inventory Visibility
description: この記事では、倉庫管理プロセス (WMS 品目) が有効になっている品目に対応した Inventory Visibility について説明します。
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762757"
---
# <a name="inventory-visibility-support-for-wms-items"></a>WMS 品目に対応した Inventory Visibility

[!include [banner](../includes/banner.md)]

この記事では、倉庫管理プロセス (WMS) が有効になっている品目に対応した Inventory Visibility について説明します。 この機能を Inventory Visibility に追加する機能は、*高度な WMS* と呼ばれています。

## <a name="wms-items"></a>WMS 品目

WMS 品目は、WMS が有効になっていて、さらに WMS が有効になっている倉庫で処理される品目です。

Microsoft Dynamics 365 Supply Chain Management の WMS および **Warehouse Management** モジュールについては、[Warehouse Management の概要](../warehousing/warehouse-management-overview.md)を参照してください。

## <a name="scope-of-the-feature"></a>機能のスコープ

Inventory Visibility の高度な WMS 機能は、手持クエリに基づく手持数量計算に焦点を当てています。 この機能は、Inventory Visibility を使用した一般的な倉庫処理活動を目的としたものではありません。 Inventory Visibility は、倉庫固有の概念をユーザーに公開するものではありません。 これらの概念の例を以下に示します。

- 引当階層
- 品目または倉庫が WMS 対応かどうか
- 単位順序グループ ID
- 倉庫固有のプロセス (出荷、積荷、ウェーブ、作業など)

Inventory Visibility は、Supply Chain Management から送信されたデータに基づいてこの情報を推測します。 WMS 固有のデータ (つまり、`WHSInventReserve` テーブルからのデータ) はユーザーに表示されません。

Inventory Visibility の高度な WMS 機能を使用すると、すべてのクエリ結果は、Supply Chain Management で直接実行されたクエリの結果と同一になります。 ただし、モバイル アプリは少し異なる計算ロジックを使用するので、Warehouse Management モバイル アプリを使用して行うクエリの結果と同一にはなりません。

## <a name="when-to-use-the-feature"></a>機能を使用する場合

次のすべての条件が満たされる場合は、Inventory Visibility に WMS 機能を使用することをお勧めします。

- Supply Chain Management のデータを Inventory Visibility と同期しています。
- Supply Chain Management で WMS を使用しています。
- ユーザーは、倉庫レベル以下のレベルで、WMS 品目の予約を行います (倉庫作業を処理しているためライセンス プレート レベルの場合など)。

他のシナリオでは、Inventory Visibility の高度な WMS 機能が有効になっているかどうかに関わらず、手持ちのクエリ結果は同一になります。 さらに、これらのシナリオでこの機能を有効にしなければ計算と間接費が減少するため、パフォーマンスが向上します。

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>Inventory Visibility のために WMS 機能を有効にする

Inventory Visibility のために WMS 機能を有効にするには、次の手順を実行します。

1. 管理者として Supply Chain Management にサインインします。
1. [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ワークスペースを開き、次の機能をこの順番で有効にします。

    1. *Inventory Visibility 統合*
    1. *Inventory Visibility で在庫品目を有効化*

1. **在庫管理 \> 設定 \> Inventory Visibility 統合パラメーター** の順に移動します。
1. **WMS 品目の有効化** タブで、**WMS 品目の有効化** オプションを *はい* に設定します。
1. Power Apps 環境にサインインし、**Inventory Visibility** を開きます。
1. **構成** ページの **機能管理** タブで、*AdvancedWHS* 機能を有効にします。
1. Supply Chain Management で、**在庫管理 \> 定期処理タスク \> Inventory Visibility 統合** の順に移動します。
1. アクション ウィンドウで **無効** を選択して、Inventory Visibility を一時的に無効にします。
1. アクション ウィンドウで **有効化** を選択して、Inventory Visibility を再度有効にします。 アドインが再読み込みされ、新しい機能が有効になります。 WMS 関連のデータが、Inventory Visibility に同期され始めます。

## <a name="query-on-hand-quantities-of-wms-items"></a>WMS 品目の手持在庫数量を照会する

WMS 品目をクエリするには、WMS 以外の品目に使用するのと同じ[アプリケーション プログラミング インターフェイス (API) およびメッセージ構文](inventory-visibility-api.md)を使用します。 品目が、WMS 品目か WMS 以外の品目であるかを指定する必要はありません。 Inventory Visibility では、保管されているデータに基づいて品目が自動的に区別されます。

WMS 品目の照会結果は、基本的に WMS 以外の品目の結果と同じです。 唯一の違いは、`fno` データ ソースからの次の物理的測定値が、Supply Chain Management の WMS ロジックに基づいて計算されることです。

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

他のすべての物理的測定値は、Inventory Visibility の WMS 機能が無効になっている場合と同じように計算されます。

WMS 品目の手持ち在庫計算の仕組みの詳細については、[Warehouse Management での引当](https://www.microsoft.com/download/details.aspx?id=43284)ホワイト ペーパーを参照してください。

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>WMS 品目の手持在庫リスト ビューおよびデータ エンティティ

**Inventory Visibility 集計のプリロード** ページには、*On-hand Index Query Preload Results* エンティティのビューが表示されます。 *Inventory summary* エンティティとは異なり、*On-hand Index Query Preload Results* エンティティは、選択した分析コードと共に製品の手持在庫リストを提供します。 Inventory Visibility により、プリロードされた集計データは 15 分おきに同期されます。

WMS 品目で Inventory Visibility を使用し、WMS 品目の手持在庫を表示する場合は、*Inventory Visibility の集計の事前読み込み* 機能を有効にすることをお勧めします ([合理化された手持在庫の事前読み込み](inventory-visibility-power-platform.md#preload-streamlined-onhand-query) も参照してください)。 Dataverse の対応するデータ エンティティは、クエリの事前読み込み結果が格納され、15 分おきに更新されます。 データ エンティティの名前は `Onhand Index Query Preload Result` です。

> [!IMPORTANT]
> Dataverse エンティティは読み取り専用です。 Inventory Visibility エンティティのデータは表示およびエクスポートできますが、**変更はできません**。

Supply Chain Management のデータ ソース (`fno`) に格納されている WMS の品目数量を変更することは禁止されています。 この動作は、Inventory Visibility の他の機能の動作に一致します。 この制限は競合を防ぐために適用されます。

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>Inventory Visibility の他の機能に対する WMS 品目の互換性

WMS 品目の [仮引当](inventory-visibility-reservations.md) と [在庫配賦](inventory-visibility-allocation.md) がサポートされます。 仮引当と配賦の算定には、WMS 関連の物理的測定値を含めることができます。

## <a name="calculate-available-to-promise-quantities"></a>納期回答可能在庫数量を計算する

このソリューションは、WMS 品目の[納期回答可能在庫 (ATP)](inventory-visibility-available-to-promise.md) を完全にサポートしています。 WMS 固有の詳細を気にせずに ATP 計算を定義できます。
