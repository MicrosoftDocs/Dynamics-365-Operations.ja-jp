---
title: ブロックされているため作業をキャンセルできない
description: ブロックされているため作業をキャンセルできない
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a24f199484c7596189b19e4cddf344e9186c6044edd2906affca9b530de44168
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722202"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>ブロックされているため作業をキャンセルできない

エラー コード: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>現象

システムは次のエラー メッセージを表示します。

> 作業 %1 は、理由タイプ %2 によってブロックされているためキャンセルできません。 キャンセルされる前に、作業のブロックを解除する必要があります。

## <a name="cause"></a>原因

作業はブロックされており、キャンセルすることができません。

**作業** ページの **一般** タブで、**ブロック** オプションが *はい* に設定されています。 この設定は、作業がブロックされていることを示します。 **ブロックの理由** タブには、作業がブロックされた理由が表示されます。

## <a name="resolution"></a>解像度

作業のブロックを解除するには、**ブロックの理由** タブを選択し、次のいずれかの手順に従います。

- **作業ブロック理由** フィールドが *未定義の理由* に設定されている場合: アクション ウィンドウの **作業** タブにある **作業** グループで、**作業のブロック解除** を選択します。
- **作業ブロック理由** フィールドが *処理中のウェーブ* に設定されている場合: アクション ウィンドウで **関連情報** タブにある **関連情報** グループで、**ウェーブ** を選択します。 **ウェーブ** ページのアクション ウィンドウで、**ウェーブ** タブにある **ウェーブ** グループで、**ウェーブ データのクリーンアップ** を選択します。

## <a name="workaround"></a>回避策

前の手順で問題が解決しなかった場合は、次の手順に従って作業をキャンセルできます。

1. **倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。
1. **作業 ID** フィールドで、キャンセルする作業の ID を指定します。現在、**作業状態** の値は、*未処理*、*進行中*、*キャンセル済*、*結合済*、または *終了済* です。
1. **OK** を選択します。
1. **はい** を選択して、作業をキャンセルすることを確認します。

詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。
