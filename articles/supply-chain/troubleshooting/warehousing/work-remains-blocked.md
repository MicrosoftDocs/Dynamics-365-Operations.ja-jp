---
title: 作業がブロックされたまま
description: 作業がブロックされたまま
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924133"
---
# <a name="work-remains-blocked"></a>作業がブロックされたまま

エラーコード: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>現象

システムは次のエラー メッセージを表示します。

> 関連付けられたサイクル %2 に状態 %3 があるため、作業 %1 はブロックされたままです。

## <a name="cause"></a>原因

次のいずれかの条件で示されているように、作業は、現在ウェーブで処理されており、ブロックを解除できません。

- **ブロックの理由** タブで、1 つ以上の明細行の **作業ブロック理由** フィールドが、*処理中のウェーブ* に設定されています。
- アクション ウィンドウの **関連情報** タブにある **関連情報** グループで **ウェーブ** を選択すると、**ウェーブステータス** フィールドが *処理中* に設定されます。

## <a name="resolution"></a>解像度

アクション ウィンドウにある **関連情報** タブの **関連情報** グループで、**ウェーブ** を選択します。 **ウェーブ** ページのアクション ウィンドウで、**ウェーブ** タブにある **ウェーブ** グループで、**ウェーブ データのクリーンアップ** を選択します。

## <a name="workaround"></a>回避策

前の手順で問題が解決しなかった場合は、次の手順に従って作業をキャンセルできます。

1. **倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。
1. **作業 ID** フィールドで、キャンセルする作業の ID を指定します。現在、**作業状態** の値は、*未処理*、*進行中*、*キャンセル済*、*結合済*、または *終了済* です。
1. **OK** を選択します。
1. **はい** を選択して、作業をキャンセルすることを確認します。

詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。
