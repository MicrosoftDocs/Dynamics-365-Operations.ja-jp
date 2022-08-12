---
title: WMS 品目に対応した Inventory Visibility
description: この記事では、倉庫管理プロセス (WMS 品目) が有効になっている品目に対応した在庫可視化について説明します。
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 54ce637d2d7b590988f7590eae5248276bcc4b96
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066613"
---
# <a name="inventory-visibility-support-for-wms-items"></a>WMS 品目に対応した Inventory Visibility

[!include [banner](../includes/banner.md)]

この記事では、倉庫管理プロセス (WMS) が有効になっている品目に対応した在庫可視化について説明します。 この機能を在庫可視化に追加する機能は、*高度な WMS* と呼ばれています。

## <a name="wms-items"></a>WMS 品目

WMS 品目は、WMS が有効になっていて、さらに WMS が有効になっている倉庫で処理される品目です。

Microsoft Dynamics 365 Supply Chain Management の WMS および **Warehouse Management** モジュールについては、[Warehouse Management の概要](../warehousing/warehouse-management-overview.md)を参照してください。

## <a name="scope-of-the-feature"></a>機能のスコープ

在庫可視化の高度な WMS 機能は、手持クエリに基づく手持数量計算に焦点を当てています。 この機能は、在庫可視化を使用した一般的な倉庫処理活動を目的としたものではありません。 在庫可視化は、倉庫固有の概念をユーザーに公開するものではありません。 これらの概念の例を以下に示します。

- 引当階層
- 品目または倉庫が WMS 対応かどうか
- 単位順序グループ ID
- 倉庫固有のプロセス (出荷、積荷、ウェーブ、作業など)

在庫可視化は、Supply Chain Management から送信されたデータに基づいてこの情報を推測します。 WMS 固有のデータ (つまり、`WHSInventReserve` テーブルからのデータ) はユーザーに表示されません。

在庫可視化の高度な WMS 機能を使用すると、すべてのクエリ結果は、Supply Chain Management で直接実行されたクエリの結果と同一になります。 ただし、モバイル アプリは少し異なる計算ロジックを使用するので、Warehouse Management モバイル アプリを使用して行うクエリの結果と同一にはなりません。

## <a name="when-to-use-the-feature"></a>機能を使用する場合

次のすべての条件が満たされる場合は、在庫可視化に高度な WMS 機能を使用することをお勧めします。

- Supply Chain Management のデータを在庫可視化と同期しています。
- Supply Chain Management で WMS を使用しています。
- ユーザーは、倉庫レベル以外のレベルで、WMS 品目の予約を行います (倉庫作業を使用している場合など)。

他のシナリオでは、在庫可視化の高度な WMS 機能が有効になっているかどうかに関わらず、手持ちのクエリ結果は同一になります。 さらに、これらのシナリオでこの機能を有効にしなければ計算と間接費が減少するため、パフォーマンスが向上します。

## <a name="enable-the-advanced-wms-feature-for-inventory-visibility"></a>在庫可視化のために高度な WMS 機能を有効にする

在庫可視化のために高度な WMS 機能を有効にするには、次の手順を実行します。

1. 管理者として Supply Chain Management にサインインします。
1. [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ワークスペースを開き、次の機能をこの順番で有効にします。

    1. *Inventory Visibility 統合*
    1. *在庫可視化で在庫品目を有効化*

1. **在庫管理 \> 設定 \> 在庫可視化統合パラメーター** の順に移動します。
1. **WMS 品目の有効化** タブで、**WMS 品目の有効化** オプションを *はい* に設定します。
1. Power Apps にサインインします。
1. **構成** ページの **機能管理** タブで、*AdvancedWHS* 機能を有効にします。
1. Supply Chain Management で、**在庫管理 \> 定期処理タスク \> 在庫可視化統合** の順に移動します。
1. アクション ウィンドウで **無効** を選択して、在庫可視化を一時的に無効にします。
1. アクション ウィンドウで **有効化** を選択して、在庫可視化を再度有効にします。 アドインが再読み込みされ、新しい機能が有効になります。 WMS 関連のデータが、在庫可視化に同期され始めます。

## <a name="query-on-hand-quantities-of-wms-items"></a>WMS 品目の手持在庫数量を照会する

WMS 品目をクエリするには、WMS 以外の品目に使用するのと同じ[アプリケーション プログラミング インターフェイス (API) およびメッセージ構文](inventory-visibility-api.md)を使用します。 品目が、WMS 品目か WMS 以外の品目であるかを指定する必要はありません。 在庫可視化では、保管されているデータに基づいて品目が自動的に区別されます。

WMS 品目の照会結果は、基本的に WMS 以外の品目の結果と同じです。 唯一の違いは、`fno` データ ソースからの次の物理的測定値が、Supply Chain Management の WMS ロジックに基づいて計算されることです。

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

他のすべての物理的測定値は、在庫可視化の高度な WMS 機能が無効になっている場合と同じように計算されます。

WMS 品目の手持ち在庫計算の仕組みの詳細については、[Warehouse Management での引当](https://www.microsoft.com/download/details.aspx?id=43284)ホワイト ペーパーを参照してください。

Dataverse にエクスポートされたデータ エンティティは、WMS 品目の数量をまだ更新できません。 データ エンティティに表示される数量は、WMS 以外の品目と、WMS ロジック (つまり、次のもの以外: `fno` データ ソースの `AvailPhysical`、`AvailOrdered`、`ReservPhysical`、`ReservOrdered`) に影響されていない数量の両方において正確です。

Supply Chain Management のデータ ソースに格納されている WMS の品目数量を変更することは禁止されています。 在庫可視化のその他の機能については、競合を防ぐためにこの制限が適用されます。

## <a name="soft-reservations-on-wms-items-in-inventory-visibility"></a>在庫可視化の WMS 品目の仮引当

一般に、WMS 品目の[仮引当](inventory-visibility-reservations.md)がサポートされています。 仮引当の算定には、WMS 関連の物理的測定値を含めることができます。 

既知の制限では、*引当可能* な計算は、現在 WMS 品目ではサポートされていません。 したがって、仮引当が発生している現在の分析コードを超える引当がある場合、*引当可能* の計算は正しくありません。 [仮引当 API](inventory-visibility-api.md#create-one-reservation-event) で **ifCheckAvailForReserv** オプションが無効になっている場合、仮引当は影響を受けません。

この制約は、仮引当 (配賦など) に基づく機能やカスタマイズにも適用されます。

## <a name="calculate-available-to-promise-quantities"></a>納期回答可能在庫数量を計算する

このソリューションは、WMS 品目の[納期回答可能在庫 (ATP)](inventory-visibility-available-to-promise.md) を完全にサポートしています。 WMS 固有の詳細を気にせずに ATP 計算を定義できます。
