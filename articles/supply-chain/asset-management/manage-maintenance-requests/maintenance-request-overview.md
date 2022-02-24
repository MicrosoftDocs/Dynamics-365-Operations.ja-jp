---
title: メンテナンス要求
description: このトピックでは、資産管理のメンテナンス要求の管理についての概要を説明します。
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e0071ae745987a1217525b2841e3320933a9242
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019632"
---
# <a name="maintenance-requests"></a>メンテナンス要求

[!include [banner](../../includes/banner.md)]

 

メンテナンス要求は、ワーク オーダーを作成せずに、資産がメンテナンスまたは修復作業を必要とする可能性があることをマネージャーまたはプランナーに通知するために作成されたメモまたは申告です。 メンテナンス要求の内容が有効と見なされる場合は、メンテナンス要求に基づいてワーク オーダーを作成することができます。

資産管理のどの資産に対しても、メンテナンス要求を作成できます。 会社のメンテナンス要求の使用方法に応じて、さまざまなタイプのメンテナンス要求を作成できます。 次にいくつか例を挙げます。

- メンテナンス要求
- 摘要
- 訂正または機能拡張
- 投資
- Depot 修復 (このタイプは、別の場所から資産を受け取りメンテナンスまたは修復作業を行い、そのジョブが完了した後に資産を返す場合に使用されます。)

## <a name="view-maintenance-requests"></a>メンテナンス要求の表示

メンテナンス要求を表示するには、**資産管理**\>**共通**\>**メンテンナンス要求**\>**すべてのメンテナンス要求**、**有効なメンテナンス要求**、または **個人用の機能的な場所のメンテナンス要求** を選択します。 各リスト ページには、メンテナンス要求に関連する情報の一部が表示されます。

![メンテナンス要求の表示](media/01-manage-maintenance-requests.png)

> [!NOTE]
> **個人用の機能的な場所のメンテナンス要求** リスト ページを使用して、作業者として関連付けられている機能的な場所、またはその機能的な場所に導入されている資産を含むメンテナンス要求のリストを表示します。 (メンテナンス作業者の機能的な場所を設定する方法については、[メンテナンス作業者および作業者グループ](../setup-for-objects/workers-and-worker-groups.md) を参照してください。)
> 
> 顧客アカウント情報は資産サービス管理 (外部メンテナンス) で使用できますが、資産管理 (内部メンテナンス) では使用できません。

レコードの詳細ビューを開くには、**すべてのメンテナンス要求** リスト ページのグリッド ビューで、**メンテナンス要求** 列のリンクを選択します。

![メンテナンス要求の詳細の表示](media/02-manage-maintenance-requests.png)

アクション ウィンドウのボタンはタブで整理されます。 次のテーブルで、資産管理に関連するボタンについて簡単に説明します。

| ボタンの名前                      | 説明 |
|----------------------------------|-------------|
| 編集                             | 選択したメンテナンス要求を編集します。 |
| 新規                              | 新しいメンテナンス要求を作成します。 |
| 消去                           | 選択したメンテナンス要求を削除します。 |
| ワーク オーダー プール                  | 選択したメンテナンス要求をワーク オーダー プールに接続します。 |
| ワーク オーダー                       | 選択したメンテナンス要求に基づいて、ワーク オーダーを作成します。 |
| 資産エラー                      | **資産エラー** をクリックすると、選択したメンテナンス要求でエラー登録を作成できます。 |
| ワーク オーダー                      | 選択したメンテナンス要求に接続されているすべてのワーク オーダーのリストを表示します。 |
| メンテナンス要求の状態の更新 | メンテナンス要求の状態を更新します。 |
| ライフサイクルの状態ログ              | 選択したメンテナンス要求のライフサイクル状態を表すログを表示します。 |
| メンテナンス要求の詳細      | 選択したメンテナンス要求の詳細を表示するレポートを印刷します。 |
| ローン資産の送信                  | 選択したメンテナンス要求で選択された資産の一時的な置換となるローン資産を選択します。 |
| ローン資産の返却                | ローン資産を返却済として登録します。 |

