---
title: 作業が未完了または不足しているため、出荷を確認できない
description: 作業が未完了または不足しているため、出荷を確認できない
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
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938505"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>作業が未完了または不足しているため、出荷を確認できない

エラーコード: WAX515

## <a name="symptoms"></a>現象

出荷を確認しようとすると、次のエラー メッセージが表示されます。

> 積荷 %1 の出荷を確定できませんでした。積荷のすべての作業を完了する必要があります。

したがって、積荷の出荷を確認できません。

## <a name="cause"></a>原因

積荷または出荷は現在、出荷確認に失敗した状態になっています。 出荷を確認する前に、少なくとも積荷の一部の作業が存在し、そのすべての作業の状態が *終了済* または *キャンセル済* である必要があります。

## <a name="resolution"></a>解像度

積荷または出荷に対して関連する販売注文または移動オーダーを確認し、関連作業がすべて完了またはキャンセルされたことを確認します。

複数のページで出荷と積荷を処理できます。 次のサブセクションでは、いくつかの例を示します。

### <a name="all-loads-page"></a>すべての積荷ページ

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を選択します。
1. アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。
1. 各作業 ID の状態を検査します。 状態が *終了済* または *キャンセル済* でない各作業 ID をフォローアップします。
1. すべての作業 ID の状態が *終了済* または *キャンセル済* である場合は、もう一度やり直して出荷を確認します。

### <a name="all-shipments-page"></a>すべての出荷ページ

1. **倉庫管理 \> 出荷 \> すべての出荷** に移動します。
1. 確認できない出荷を選択します。
1. アクション ウィンドウの **出荷** タブの、**作業** グループで、**作業詳細** を選択します。
1. 各作業 ID の状態を検査します。 状態が *終了済* または *キャンセル済* でない各作業 ID をフォローアップします。
1. すべての作業 ID の状態が *終了済* または *キャンセル済* である場合は、もう一度やり直して出荷を確認します。

### <a name="all-work-page"></a>すべての作業ページ

1. **倉庫管理 \> 作業 \> すべての作業** の順に移動します。
1. 出荷を確認できない注文番号の作業を選択します。
1. アクション ウィンドウの **出荷** タブの、**出荷** グループで、**出荷の確認** を選択します。
1. 各作業 ID の状態を検査します。 状態が *終了済* または *キャンセル済* でない各作業 ID をフォローアップします。
1. すべての作業 ID の状態が *終了済* または *キャンセル済* である場合は、もう一度やり直して出荷を確認します。
