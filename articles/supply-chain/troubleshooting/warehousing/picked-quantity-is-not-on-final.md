---
title: 品目がピッキングされていないため、出荷を確認できない
description: 品目がピッキングされていないため、出荷を確認できない
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7b57d3151852c9a2880185b7d9414e4246b7efb6429fcfce04c7cdae4ee00e37
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760927"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>品目がピッキングされていないため、出荷を確認できない

エラー コード: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>現象

出荷を確認しようとすると、次のエラー メッセージが表示されます。

> 積荷 %1 に必要な一部の品目がまだピッキングされておらず、最終出荷場所に移動されていません。

したがって、積荷の出荷を確認できません。

## <a name="cause"></a>原因

次のいずれかの条件が存在する可能性があるため、現在の状態では積荷または出荷を確認できません:

- 関連する作業がまだ選択されていないので、最終的な出荷場所に移動されていません。
- 作業のピッキング済数量が、積荷明細行で作成された作業数量と一致しません。
- ウェーブ テンプレートのコンテナー詰めの使用中に、梱包場所を最終的な出荷場所として使用して、場所のディレクティブが構成されました。

## <a name="resolution"></a>解決策

積荷または出荷は現在、出荷確認に失敗した状態になっています。 この問題を解決するには、次のいずれかのタスクを実行します。

- 積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。
- 最終的な出荷場所として梱包場所を使用するように作成した作業 ID をキャンセルし、場所のディレクティブを変更し、積荷を再リリースします。

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します

次の手順を使用して積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を選択します。
1. **積荷明細行** クイックタブで、積荷明細行を選択します。
1. **作業作成数量** フィールドの値を記録します。
1. アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。
1. 作業が最後の出荷場所で完了し、作業のピッキング済数量が積荷明細行で作成された作業数量と一致していることを確認します。
1. すべての積荷明細行に対してこの手順を繰り返して、すべての基準が満たされていることを確認します。

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>最終的な出荷場所として梱包場所を使用するように作成した作業 ID をキャンセルし、場所のディレクティブを変更し、積荷を再リリースする

次の手順を使用して、梱包場所を自動コンテナ詰めが設定された最終的な配置場所とする作業 ID をキャンセルします。

1. **倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。
1. **作業のキャンセル** ダイアログ ボックスが開きます。 **作業 ID** フィールドで、キャンセルする作業の ID を指定します。 選択した作業 ID は、**作業状態** の値が *開く*、*処理中*、*処理済*、*結合済*、または *クローズ済* であることが必要です。
1. **OK** を選択します。
1. **はい** を選択して、作業をキャンセルすることを確認します。
1. 必要に応じて他の作業 ID に対して、この手順を繰り返します。

詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。

次の手順に従って、自動コンテナ詰めがウェーブ テンプレートに設定されているときに、梱包場所を最終的な出荷場所として使用しないよう、場所のディレクティブを再構成します。

1. **倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。
1. **ワーク オーダー タイプ** フィールドで、*販売注文* を選択します。
1. 自動コンテナ詰めに使用している場所のディレクティブを選択します。
1. **場所ディレクティブ アクション** クイックタブ ツールバーで、**クエリの編集** を選択します。
1. クエリ エディター ダイアログボックスの **範囲** タブで、**フィールド** が *場所プロファイル* に設定されている行を検索し、その行の **基準** フィールドが **場所タイプ** が *梱包* である場所プロファイルに設定されていないか確認します。 **基準** フィールドを調整し、最終的な配置場所を修正します。

次の手順を使用して積荷を再リリースし、最終的な出荷場所が正しい作業 ID を作成します。

1. **倉庫管理 \> 積荷 \> 積荷計画ワークベンチ** に移動します。
1. **積荷** セクションで、リリースする必要がある積荷を検索します。
1. **積荷** セクションのツールバーで、**リリース \> 倉庫へのリリース** を選択し、選択した積荷を倉庫にリリースします。
1. 必要に応じて他の積荷に対して、この手順を繰り返します。
