---
title: 最後の終了した作業明細行をプットにする必要がある
description: 最後の終了した作業明細行をプットにする必要がある
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924378"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>最後の終了した作業明細行をプットにする必要がある

エラーコード: WAX1285

## <a name="symptoms"></a>現象

システムは次のエラー メッセージを表示します。

> 最後の終了した作業明細行はプットにする必要があります。

## <a name="cause"></a>原因

現在の状態では、作業をキャンセルできません。

最後の作業明細行では、**作業状態** フィールドは *クローズ済* に設定されていますが、**作業タイプ** フィールドは *プット* に設定されていません。

## <a name="resolution"></a>解像度

作業をキャンセルするには、これらの手順に従います。

1. **倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。
1. **作業 ID** フィールドで、キャンセルする作業の ID を指定します。
1. **OK** を選択します。
1. **はい** を選択して、作業をキャンセルすることを確認します。

詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。
